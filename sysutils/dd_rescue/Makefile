# Created by: MANTANI Nobutaka <nobutaka@FreeBSD.org>
# $FreeBSD$

PORTNAME=	dd_rescue
PORTVERSION=	1.46
CATEGORIES=	sysutils
MASTER_SITES=	http://www.garloff.de/kurt/linux/ddrescue/ \
		http://fossies.org/unix/privat/

MAINTAINER=	nobutaka@FreeBSD.org
COMMENT=	dd tool suitable for rescuing data from a medium with errors

LICENSE=	GPLv2
LICENSE_FILE=	${WRKSRC}/COPYING

USES=		gmake
USE_CSTD=	gnu89
USE_AUTOTOOLS=	autoconf autoheader

WRKSRC=		${WRKDIR}/${PORTNAME}
ALL_TARGET=	default

OPTIONS_DEFINE=	DOCS

.include <bsd.port.options.mk>
.include <bsd.port.pre.mk>

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/dd_rescue ${STAGEDIR}${PREFIX}/bin
	${INSTALL_PROGRAM} ${WRKSRC}/libddr_hash.so ${STAGEDIR}${PREFIX}/lib
	${INSTALL_PROGRAM} ${WRKSRC}/libddr_null.so ${STAGEDIR}${PREFIX}/lib
	${INSTALL_MAN} ${WRKSRC}/dd_rescue.1 ${STAGEDIR}${PREFIX}/man/man1
.if ${PORT_OPTIONS:MDOCS}
	${MKDIR} ${STAGEDIR}${DOCSDIR}
	${INSTALL_DATA}	${WRKSRC}/README.dd_rescue ${STAGEDIR}${DOCSDIR}
.endif

.include <bsd.port.post.mk>
