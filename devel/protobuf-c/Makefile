# Created by: Aaron Hurt <ahurt@anbcs.com>
# $FreeBSD$

PORTNAME=		protobuf-c
PORTVERSION=		1.1.1
DISTVERSIONPREFIX=	v
CATEGORIES=		devel

MAINTAINER=	truckman@FreeBSD.org
COMMENT=	Code generator and libraries to use Protocol Buffers from pure C

LICENSE=	BSD2CLAUSE
LICENSE_FILE=	${WRKSRC}/LICENSE

LIB_DEPENDS=	libprotobuf.so:${PORTSDIR}/devel/protobuf

USES=		autoreconf gmake libtool pkgconfig
GNU_CONFIGURE=	yes
USE_GITHUB=	yes
USE_LDCONFIG=	yes

CPPFLAGS+=	-I${LOCALBASE}/include
LDFLAGS+=	-L${LOCALBASE}/lib

OPTIONS_DEFINE=	DOXYGEN
OPTIONS_DEFAULT=	DOXYGEN

PORTDOCS=	*

ALL_TARGET=	all
INSTALL_TARGET=	install-strip
DOXYGEN_BUILD_DEPENDS=	doxygen:${PORTSDIR}/devel/doxygen
DOXYGEN_ALL_TARGET=	html-local

.include <bsd.port.options.mk>

.if ${PORT_OPTIONS:MDOXYGEN}
post-install:
	@${MKDIR} ${STAGEDIR}${DOCSDIR}/html
	${INSTALL_DATA} ${WRKSRC}/html/* ${STAGEDIR}${DOCSDIR}/html
.endif

tests: build
	@(cd ${WRKSRC} && ${SETENV} ${MAKE_ENV} ${MAKE} ${MAKE_FLAGS} ${MAKEFILE} ${MAKE_ARGS} check)

.include <bsd.port.mk>
