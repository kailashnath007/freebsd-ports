# Created by: Michael Johnson <ahze@FreeBSD.org>
# $FreeBSD$

PORTREVISION=	2
PKGNAMEPREFIX=	p5-

COMMENT=	Perl API for QDBM

SLAVEPORT=	perl
USES=		perl5 shebangfix

MASTERDIR=	${.CURDIR}/../../databases/qdbm
WRKSRC=		${WRKDIR}/${PORTNAME}-${PORTVERSION}/perl
PLIST=		${.CURDIR}/pkg-plist
DESCR=		${.CURDIR}/pkg-descr
PATCHDIR=	${.CURDIR}/files

SHEBANG_FILES=	mypldoc curia/plcrtest depot/pldptest villa/plvltest

MAKE_JOBS_UNSAFE=	yes

MAKE_ARGS=	LD=${CC}

.include "${MASTERDIR}/Makefile"
