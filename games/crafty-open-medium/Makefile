# Created by: Stefan Eggers <seggers@semyam.dinoco.de>
# $FreeBSD$

PORTNAME=	crafty-open-medium
PORTVERSION=	20070909
PORTREVISION=	2
CATEGORIES=	games
MASTER_SITES=	LOCAL/dd/crafty
DISTNAME=	medium

MAINTAINER=	ports@FreeBSD.org
COMMENT=	The medium opening book (about 1.9 MByte) for crafty

BUILD_DEPENDS=	crafty:${PORTSDIR}/games/crafty
RUN_DEPENDS=	crafty:${PORTSDIR}/games/crafty

DIST_SUBDIR=	crafty
USES=		zip
NO_WRKSUBDIR=	yes
CONFLICTS=	crafty-open-enormous-* crafty-open-large-* crafty-open-default-*

do-build:
	@${ECHO_MSG} '================================================================'
	@${ECHO_MSG} 'Ignore warnings about illegal moves.  These warnings are normal.'
	@${ECHO_MSG} '================================================================'
	(${CHOWN} nobody ${WRKDIR}; cd ${WRKDIR}; crafty <${FILESDIR}/book-building)

do-install:
	@${MKDIR} ${STAGEDIR}${PREFIX}/lib/crafty
	${INSTALL_DATA} ${WRKDIR}/book.bin \
		${STAGEDIR}${PREFIX}/lib/crafty/book.bin
	${CHOWN} nobody:nogroup ${STAGEDIR}${PREFIX}/lib/crafty/book.bin
	${CHMOD} 664 ${STAGEDIR}${PREFIX}/lib/crafty/book.bin

.include <bsd.port.mk>
